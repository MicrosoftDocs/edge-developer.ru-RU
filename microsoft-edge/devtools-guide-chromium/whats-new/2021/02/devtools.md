---
description: Поддержка отладки для CSS Flexbox, отображение на веб-странице над головой производительности, выпуск обновлений инструментов и другие
title: Новые возможности в DevTools (Microsoft Edge 90)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 4222bcf7284b69269691ec9fb78094e5efb95793
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408561"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-90"></a><span data-ttu-id="16ced-104">Что нового в DevTools (Microsoft Edge 90)</span><span class="sxs-lookup"><span data-stu-id="16ced-104">What's New In DevTools (Microsoft Edge 90)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="group-tools-together-in-focus-mode"></a><span data-ttu-id="16ced-105">Групповые инструменты вместе в режиме Фокус</span><span class="sxs-lookup"><span data-stu-id="16ced-105">Group tools together in Focus Mode</span></span>  

<!-- Title: Grouping the tools in Focus Mode  -->  
<!-- Subtitle: Organize your favorite tools into groups with the new Focus Mode UI.  -->  

<span data-ttu-id="16ced-106">Focus Mode — это экспериментальный интерфейс, который позволяет сгруппировать различные инструменты вместе на основе собственных сценариев отладки.</span><span class="sxs-lookup"><span data-stu-id="16ced-106">Focus Mode is an experimental interface that allows you to group different tools together based on your own debugging scenarios.</span></span>  <span data-ttu-id="16ced-107">Новая **планка действий,** отображаемая слева, включает предопределяющие группы инструментов, такие как **Layout** и **Debugging.**</span><span class="sxs-lookup"><span data-stu-id="16ced-107">The new **Activity Bar** displayed on the left includes predefined tool groups such as **Layout** and **Debugging**.</span></span>  <span data-ttu-id="16ced-108">Чтобы настроить каждую группу инструментов, закройте инструменты значком **Close** \( \) или добавьте новые средства с значком `X` More **tools** `+` \( \) .</span><span class="sxs-lookup"><span data-stu-id="16ced-108">To customize each tool group, close tools with the **Close** \(`X`\) icon or add new tools with the **More tools** \(`+`\) icon.</span></span>  

<span data-ttu-id="16ced-109">Чтобы включить эксперимент, перейдите к включаем экспериментальные функции и выберите контрольные ящики рядом с режимом Фокус и **Инструменты DevTools** и **включить +** меню вкладок кнопки, чтобы открыть дополнительные средства . [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="16ced-109">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="16ced-110">Дополнительные сведения об этой функции или комментарии с вопросами и идеями перейдите к [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="16ced-110">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode.msft.png" alt-text="Отображение панели действий" lightbox="../../media/2021/02/focus-mode.msft.png":::
   <span data-ttu-id="16ced-112">Отображение **панели действий**</span><span class="sxs-lookup"><span data-stu-id="16ced-112">Display the **Activity Bar**</span></span>  
:::image-end:::  

## <a name="learn-about-devtools-with-informative-tooltips"></a><span data-ttu-id="16ced-113">Узнайте о DevTools с помощью информационных инструментов</span><span class="sxs-lookup"><span data-stu-id="16ced-113">Learn about DevTools with informative tooltips</span></span>  

<!-- Title: DevTools Tooltips  -->  
<!-- Subtitle: Learn more about how to use DevTools with informative DevTools tooltips.  -->  

<span data-ttu-id="16ced-114">Функция Tooltips DevTools поможет вам узнать обо всех различных средствах и стеколах.</span><span class="sxs-lookup"><span data-stu-id="16ced-114">The DevTools Tooltips feature helps you learn about all the different tools and panes.</span></span>  <span data-ttu-id="16ced-115">Выберите значок Справка \( \) в нижней части панели действий, чтобы перегнастить инструменты `?` в DevTools. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="16ced-115">Choose the Help \(`?`\) icon at the bottom of the **Activity Bar** to toggle tooltips in the DevTools.</span></span>  <span data-ttu-id="16ced-116">Когда используются инструменты, наведите курсор на каждый из описанных областей DevTools, чтобы узнать больше о том, как использовать средство.</span><span class="sxs-lookup"><span data-stu-id="16ced-116">When tooltips are on, hover over each outlined region of DevTools to learn more about how to use the tool.</span></span>  <span data-ttu-id="16ced-117">Чтобы включить эксперимент, перейдите к включаем экспериментальные функции и выберите контрольные ящики рядом с режимом Фокус и **Инструменты DevTools** и **включить +** меню вкладок кнопки, чтобы открыть дополнительные средства . [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="16ced-117">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkboxes next to **Focus Mode and DevTools Tooltips** and **Enable + button tab menus to open more tools**.</span></span>  <span data-ttu-id="16ced-118">Дополнительные сведения об этой функции или комментарии с вопросами и идеями перейдите к [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span><span class="sxs-lookup"><span data-stu-id="16ced-118">For more information about this feature or to comment with questions and ideas, navigate to [DevTools: Focus Mode UI][GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer].</span></span>  

:::image type="complex" source="../../media/2021/02/focus-mode-and-tooltips-help.msft.png" alt-text="Выберите значок Справка (?) в панели действий для отображения наборов инструментов" lightbox="../../media/2021/02/focus-mode-and-tooltips-help.msft.png":::
   <span data-ttu-id="16ced-120">Выберите значок Справка `?` \( \) в панели **действий для** отображения наборов инструментов</span><span class="sxs-lookup"><span data-stu-id="16ced-120">Choose the Help \(`?`\) icon in the **Activity Bar** to display tooltips</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="16ced-121">Настройка ярлыков клавиатуры в параметрах</span><span class="sxs-lookup"><span data-stu-id="16ced-121">Customize keyboard shortcuts in Settings</span></span>  

<!-- Title: Change keyboard shortcuts in Settings  -->  
<!-- TODO:  Rachel's feedback is about the fact that this experimental feature is turned on by default, may have separate section in What's New for experimental features)  -->  
<!-- Subtitle: Make DevTools work better for you by creating new keyboard shortcuts for any action in the DevTools.  -->  

<span data-ttu-id="16ced-122">Теперь можно настроить ярлык клавиатуры для любых действий в DevTools.</span><span class="sxs-lookup"><span data-stu-id="16ced-122">You may now customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="16ced-123">Чтобы изменить ярлык клавиатуры, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="16ced-123">To edit a keyboard shortcut, complete the following actions.</span></span>  

1.  <span data-ttu-id="16ced-124">Откройте DevTools и выберите **ярлыки**  >  **Параметры.**</span><span class="sxs-lookup"><span data-stu-id="16ced-124">Open the DevTools, and then choose **Settings** > **Shortcuts**.</span></span>  
1.  <span data-ttu-id="16ced-125">Выберите действие, необходимое для настройки.</span><span class="sxs-lookup"><span data-stu-id="16ced-125">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="16ced-126">Выбор редактирования \.</span><span class="sxs-lookup"><span data-stu-id="16ced-126">Choose the Edit \(</span></span>![Изменение значка ярлыка клавиатуры](../../media/2021/02/edit-keyboard-shortcut-icon.msft.png)<span data-ttu-id="16ced-128">\) значок.</span><span class="sxs-lookup"><span data-stu-id="16ced-128">\) icon.</span></span>  
1.  <span data-ttu-id="16ced-129">Выберите клавиши, которые необходимо привязать к действию.</span><span class="sxs-lookup"><span data-stu-id="16ced-129">Select the keys you want to bind to the action.</span></span>  
1.  <span data-ttu-id="16ced-130">Выбор контрольного знака \.</span><span class="sxs-lookup"><span data-stu-id="16ced-130">Choose the checkmark \(</span></span>![Значок ярлыка клавиатуры checkmark](../../media/2021/02/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="16ced-132">\) значок.</span><span class="sxs-lookup"><span data-stu-id="16ced-132">\) icon.</span></span>  
    
<span data-ttu-id="16ced-133">Дополнительные сведения о настройке и редактировании ярлыков перейдите к настройкам клавиш в [Microsoft Edge DevTools.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="16ced-133">For more information about customizing and editing shortcuts, navigate to [Customize keyboard shortcuts in the Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="16ced-134">Чтобы просмотреть обновления в режиме реального времени по этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="16ced-134">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png" alt-text="Настройка ярлыков клавиатуры в параметрах DevTools на ярлыках с помощью ярлыка в режиме редактирования" lightbox="../../media/2021/02/custom-shortcut-pause-script-checkmark.msft.png":::
   <span data-ttu-id="16ced-136">Настройка ярлыков клавиатуры в [параметрах DevTools][DevtoolsCustomizeIndexSettings] на ярлыках с помощью ярлыка в режиме редактирования</span><span class="sxs-lookup"><span data-stu-id="16ced-136">Customize keyboard shortcuts in the [DevTools Settings][DevtoolsCustomizeIndexSettings] on Shortcuts with a shortcut in edit mode</span></span>  
:::image-end:::  

## <a name="microsoft-edge-devtools-for-visual-studio-code-extension-update-114"></a><span data-ttu-id="16ced-137">Microsoft Edge DevTools для Visual Studio обновления расширения кода 1.1.4</span><span class="sxs-lookup"><span data-stu-id="16ced-137">Microsoft Edge DevTools for Visual Studio Code extension update 1.1.4</span></span>  

<!-- Title: Edge Devtools for Visual Studio code extension update 1.1.4  -->  
<!-- Subtitle: Latest changes including a favicon is displayed next to each of the instances and console messages from the browser are displayed in the console of Visual Studio Code.  -->  

<span data-ttu-id="16ced-138">В [microsoft Edge Developer Tools для Visual Studio][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] версии 1.1.4 для Microsoft Visual Studio Code теперь отображается февикон рядом с каждым экземпляром DevTools.</span><span class="sxs-lookup"><span data-stu-id="16ced-138">The [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.4 for Microsoft Visual Studio Code now displays a favicon next to each of the DevTools instances.</span></span>  <span data-ttu-id="16ced-139">Консольные сообщения от Microsoft Edge теперь отображаются в **консоли DevTools** в статье **Output** of Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="16ced-139">Console messages from Microsoft Edge now display in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  <span data-ttu-id="16ced-140">Microsoft Visual Studio обновления кода автоматически.</span><span class="sxs-lookup"><span data-stu-id="16ced-140">Microsoft Visual Studio Code updates extensions automatically.</span></span>  <span data-ttu-id="16ced-141">Чтобы вручную обновить версию 1.1.4, перейдите к [обновлению расширения вручную.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]</span><span class="sxs-lookup"><span data-stu-id="16ced-141">To manually update to version 1.1.4, navigate to [Update an extension manually][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually].</span></span>  <span data-ttu-id="16ced-142">Вы можете файл проблемы и внести свой вклад в расширение [на vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub репо.</span><span class="sxs-lookup"><span data-stu-id="16ced-142">You may file issues and contribute to the extension on the [vscode-edge-devtools][GithubMicrosoftVscodeEdgeDevtools] GitHub repo.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="16ced-143">На следующем рисунке отображаются сообщения с веб-страницы примера, зарегистрированной **в** консоли в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="16ced-143">The following figure displays messages from an example webpage logged in the **Console** tool in Microsoft Edge.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="16ced-144">На следующем рисунке отображаются те же сообщения с веб-страницы примера, зарегистрированной в **консоли DevTools** в **статье Output** of Microsoft Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="16ced-144">The following figure displays the same messages from the example webpage logged in the **DevTools Console** under **Output** of Microsoft Visual Studio Code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png" alt-text="Отображение сообщения в консоли в Microsoft Edge DevTools" lightbox="../../media/2021/02/visual-studio-code-extension-log-microsoft-edge.msft.png":::
         <span data-ttu-id="16ced-146">Отображение сообщения в консоли в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="16ced-146">Display a message in Console in Microsoft Edge DevTools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png" alt-text="Отображение того же сообщения в консоли DevTools в статье Output of Microsoft Visual Studio Code" lightbox="../../media/2021/02/visual-studio-code-extension-log-editor.msft.png":::
         <span data-ttu-id="16ced-148">Отображение того же сообщения в консоли DevTools в статье Output of Microsoft Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="16ced-148">Display the same message in the DevTools Console under Output of Microsoft Visual Studio Code</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-flexbox-editing-with-visual-flexbox-editor-and-multiple-overlays"></a><span data-ttu-id="16ced-149">Улучшенное редактирование flexbox CSS с помощью визуального редактора flexbox и нескольких накладок</span><span class="sxs-lookup"><span data-stu-id="16ced-149">Improved CSS flexbox editing with visual flexbox editor and multiple overlays</span></span>  

<!-- Title: Try different CSS flexbox layouts with the visual flexbox editor  -->  
<!-- Subtitle: In the Styles pane, choose the icon that appears next to display: flex to try different layout properties for flex containers.  -->  

<span data-ttu-id="16ced-150">DevTools теперь имеет выделенные средства отладки flexbox CSS.</span><span class="sxs-lookup"><span data-stu-id="16ced-150">DevTools now has dedicated CSS flexbox debugging tools.</span></span>  <span data-ttu-id="16ced-151">Если стиль CSS применяется к элементу HTML, значок отображается рядом с этим элементом в `display: flex` `display: inline-flex` `flex` **средстве Elements.**</span><span class="sxs-lookup"><span data-stu-id="16ced-151">If the `display: flex` or `display: inline-flex` CSS style is applied to an HTML element, a `flex` icon displays next to that element in the **Elements** tool.</span></span>  <span data-ttu-id="16ced-152">Чтобы отобразить на веб-странице наложение flex \(или скрыть\) выберите `flex` значок.</span><span class="sxs-lookup"><span data-stu-id="16ced-152">To display \(or hide\) a flex overlay on the webpage, choose the `flex` icon.</span></span>  <span data-ttu-id="16ced-153">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1166710][CR1166710] и [1175699][CR1175699].</span><span class="sxs-lookup"><span data-stu-id="16ced-153">To review the history of this feature in the Chromium open-source project, navigate to Issues [1166710][CR1166710] and [1175699][CR1175699].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="16ced-154">Чтобы открыть **редактор Flexbox,** перейдите на области **Стилей** и выберите новый значок рядом с `display: flex` `display: inline-flex` стилем или стилем.</span><span class="sxs-lookup"><span data-stu-id="16ced-154">To open the **Flexbox** editor, navigate to the **Styles** pane and choose the new icon next to the `display: flex` or `display: inline-flex` style.</span></span>  <span data-ttu-id="16ced-155">Редактор **Flexbox** предоставляет быстрый способ редактирования свойств flexbox.</span><span class="sxs-lookup"><span data-stu-id="16ced-155">The **Flexbox** editor provides a quick way to edit the flexbox properties.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="16ced-156">Кроме того, раздел **Flexbox** в области **Макет** отображает все элементы flexbox на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="16ced-156">In addition, the **Flexbox** section in the **Layout** pane displays all of the flexbox elements on the webpage.</span></span>  <span data-ttu-id="16ced-157">Можно перенакладку каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="16ced-157">You may toggle the overlay of each element.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-styles-display-flex-window.msft.png" alt-text="Средства отладки flexbox CSS" lightbox="../../media/2021/02/elements-styles-display-flex-window.msft.png":::
         <span data-ttu-id="16ced-159">Средства отладки flexbox CSS</span><span class="sxs-lookup"><span data-stu-id="16ced-159">CSS flexbox debugging tools</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png" alt-text="Раздел Flexbox в области Макет" lightbox="../../media/2021/02/elements-layout-flexbox-flexbox-overlays.msft.png":::
         <span data-ttu-id="16ced-161">**Раздел Flexbox** в области **Макет**</span><span class="sxs-lookup"><span data-stu-id="16ced-161">**Flexbox** section in the **Layout** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="keyboard-navigation-improvements-for-network-requests"></a><span data-ttu-id="16ced-162">Улучшения навигации по клавиатуре для сетевых запросов</span><span class="sxs-lookup"><span data-stu-id="16ced-162">Keyboard navigation improvements for network requests</span></span>  

<!-- Title: Navigate the request initiator chain in the Network tool with the keyboard  -->  
<!-- Subtitle: The Initiator pane may now be expanded or collapsed with the arrow keys.  -->  

<span data-ttu-id="16ced-163">Ранее вы не могли расширить или свернуть цепочку запросов с помощью \*\*\*\* клавиш стрелки на клавиатуре в области Инициатор, в отличие от DOM в **инструменте Elements.**</span><span class="sxs-lookup"><span data-stu-id="16ced-163">Previously, you were not able to expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane, unlike the DOM in the **Elements** tool.</span></span>  <span data-ttu-id="16ced-164">При выборе сетевого запроса в средстве **Network** в области Инициатор отображает цепочку запросов, которые инициировали выбранный в настоящее время запрос. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="16ced-164">When a network request is selected in the **Network** tool, the **Initiator** pane displays the chain of requests that initiated the currently selected request.</span></span>  

<span data-ttu-id="16ced-165">В microsoft Edge версии 90 можно расширить или свернуть цепочку запросов с помощью клавиш стрелки на клавиатуре в области **Инициатор.**</span><span class="sxs-lookup"><span data-stu-id="16ced-165">In Microsoft Edge version 90, you may expand or collapse the chain of requests using the arrow keys on the keyboard in the **Initiator** pane.</span></span>  <span data-ttu-id="16ced-166">Фокусный запрос сети в цепочке также теперь выделен.</span><span class="sxs-lookup"><span data-stu-id="16ced-166">The focused network request in the chain is also now highlighted.</span></span>  <span data-ttu-id="16ced-167">Чтобы узнать больше о инициаторах в средстве **Network,** перейдите к [инициаторам отображения и зависимостей.][DevtoolsNetworkReferenceDisplayInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="16ced-167">To learn more about initiators in the **Network** tool, navigate to [Display initiators and dependencies][DevtoolsNetworkReferenceDisplayInitiatorsDependencies].</span></span>  <span data-ttu-id="16ced-168">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [1158276][CR1158276] и [1160637][CR1160637].</span><span class="sxs-lookup"><span data-stu-id="16ced-168">To review the history of this feature in the Chromium open-source project, navigate to Issues [1158276][CR1158276] and [1160637][CR1160637].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain.msft.png" alt-text="Выберите запрос Сети и выберите области инициатора" lightbox="../../media/2021/02/network-request-initiator-chain.msft.png":::
         <span data-ttu-id="16ced-170">Выберите запрос Сети и выберите области **инициатора**</span><span class="sxs-lookup"><span data-stu-id="16ced-170">Choose a Network request and choose the **Initiator** pane</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png" alt-text="Расширение или свернуть цепочку инициатора запроса и следовать выделенной строке" lightbox="../../media/2021/02/network-request-initiator-chain-right-arrow-down-twice-down-arrow-thrice.msft.png":::
         <span data-ttu-id="16ced-172">Расширение или свернуть цепочку инициатора запроса и следовать выделенной строке</span><span class="sxs-lookup"><span data-stu-id="16ced-172">Expand or collapse the request initiator chain and follow the highlighted row</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="filtering-in-the-console-is-more-consistent"></a><span data-ttu-id="16ced-173">Фильтрация в консоли более согласована</span><span class="sxs-lookup"><span data-stu-id="16ced-173">Filtering in the Console is more consistent</span></span>  

<!-- Title: Console improvements make filtering more consistent  -->  
<!-- Subtitle: The Log Levels dropdown is more clearly disabled when using filters in the Console sidebar.  -->  

<span data-ttu-id="16ced-174">При фильтрации с [боковой панелью][DevtoolsConsoleReferenceOpenConsoleSidebar]консоли [][DevtoolsConsoleReferenceFilterByLogLevel] фильтры в отсеве уровней журналов недоступны.</span><span class="sxs-lookup"><span data-stu-id="16ced-174">While you filter with the [Console Sidebar][DevtoolsConsoleReferenceOpenConsoleSidebar], the filters in the [Log Levels][DevtoolsConsoleReferenceFilterByLogLevel] dropdown are not available.</span></span>  <span data-ttu-id="16ced-175">Ранее **отсев уровней** журналов выделялся при наведении на \*\*\*\* него, даже если был выбран фильтр из боковой панели консоли.</span><span class="sxs-lookup"><span data-stu-id="16ced-175">Previously, the **Log Levels** dropdown highlighted when you hovered on it, even while a filter from the **Console Sidebar** was chosen.</span></span>  <span data-ttu-id="16ced-176">В Microsoft Edge версии 90 отсев уровней журналов больше не выделяется при наведении на нем при выборе фильтра из боковой панели консоли. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="16ced-176">In Microsoft Edge version 90, the **Log Levels** dropdown no longer highlights when you hover on it while a filter from the **Console Sidebar** is chosen.</span></span>  <span data-ttu-id="16ced-177">Чтобы узнать больше о фильтрации в **консоли,** перейдите к [фильтрации сообщений][DevtoolsConsoleReferenceFilterMessages].</span><span class="sxs-lookup"><span data-stu-id="16ced-177">To learn more about filtering in the **Console**, navigate to [Filter Messages][DevtoolsConsoleReferenceFilterMessages].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-old.msft.png" alt-text="Ранее, если вы откроете боковую панель консоли и наведите курсор на уровнях по умолчанию, она была выделена" lightbox="../../media/2021/02/console-sidebar-default-levels-old.msft.png":::
         <span data-ttu-id="16ced-179">Ранее, если вы откроете **боковую** панель консоли и наведите курсор на уровнях **по** умолчанию, она была выделена</span><span class="sxs-lookup"><span data-stu-id="16ced-179">Previously, if you open the **Console sidebar** and hover on **Default levels** it was highlighted</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/console-sidebar-default-levels-new.msft.png" alt-text="Начиная с Microsoft Edge 90, если выбрать боковую панель консоли и наведении на уровнях по умолчанию, она не выделяется" lightbox="../../media/2021/02/console-sidebar-default-levels-new.msft.png":::
         <span data-ttu-id="16ced-181">Начиная с Microsoft Edge 90, если выбрать боковую панель **консоли** и наведении на уровнях по **умолчанию,** она не выделяется</span><span class="sxs-lookup"><span data-stu-id="16ced-181">Starting in Microsoft Edge 90, if you choose the **Console sidebar** and hover on **Default levels**, it does not highlight</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="16ced-182">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="16ced-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="the-console-now-escapes-double-quote-characters"></a><span data-ttu-id="16ced-183">Консоль теперь избегает символов двойной кавычка</span><span class="sxs-lookup"><span data-stu-id="16ced-183">The Console now escapes double quote characters</span></span>  

<span data-ttu-id="16ced-184">Ранее консоль не **выводит** допустимые двойные кавычка `"` \( \) символов в строках JavaScript.</span><span class="sxs-lookup"><span data-stu-id="16ced-184">Previously, the **Console** did not output valid double quote \(`"`\) characters in JavaScript strings.</span></span>  <span data-ttu-id="16ced-185">Начиная с microsoft Edge версии \*\*\*\* 90, консоль выводит строки JavaScript с использованием избежавных двойных кавычков `"` \( \) символов.</span><span class="sxs-lookup"><span data-stu-id="16ced-185">Starting in Microsoft Edge version 90, the **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters.</span></span>  <span data-ttu-id="16ced-186">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1178530][CR1178530].</span><span class="sxs-lookup"><span data-stu-id="16ced-186">To review the history of this feature in the Chromium open-source project, navigate to Issue [1178530][CR1178530].</span></span>  

:::image type="complex" source="../../media/2021/02/console-string-formatted-double-quotes.msft.png" alt-text="Консоль выводит строки JavaScript с помощью сбежавных символов двойной &#0022;" lightbox="../../media/2021/02/console-string-formatted-double-quotes.msft.png":::
   <span data-ttu-id="16ced-188">Консоль **выводит** строки JavaScript с помощью сбежавных символов двойной `"` цитаты \( \)</span><span class="sxs-lookup"><span data-stu-id="16ced-188">The **Console** outputs JavaScript strings using escaped double quote \(`"`\) characters</span></span>  
:::image-end:::  

### <a name="emulate-the-css-color-gamut-media-feature"></a><span data-ttu-id="16ced-189">Эмулировать функцию CSS цветовой гаммы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="16ced-189">Emulate the CSS color-gamut media feature</span></span>  

<span data-ttu-id="16ced-190">Запрос [мультимедиа с цветовой][ChromestatusFeature5354410980933632] гаммой эмулирует примерный диапазон цветов, поддерживаемых браузером, и тестируемого устройства.</span><span class="sxs-lookup"><span data-stu-id="16ced-190">The [color-gamut][ChromestatusFeature5354410980933632] media query emulates the approximate range of colors supported by the browser and the device you are testing.</span></span>  <span data-ttu-id="16ced-191">Выпадательная информация под **эмулировать цветовую гамму CSS-мультимедиа** содержит цветовые пространства, которые могут эмулировать DevTools.</span><span class="sxs-lookup"><span data-stu-id="16ced-191">The dropdown under **Emulate CSS media feature color-gamut** contains color spaces that DevTools may emulate.</span></span>  <span data-ttu-id="16ced-192">Например, чтобы вызвать запрос `color-gamut: p3` мультимедиа, выберите **цветовую гамму: p3** из отсеки.</span><span class="sxs-lookup"><span data-stu-id="16ced-192">For example, to trigger a `color-gamut: p3` media query, choose **color-gamut: p3** from the dropdown.</span></span>  

<span data-ttu-id="16ced-193">Чтобы подражать функции CSS цветовой гаммы мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="16ced-193">To emulate the CSS color-gamut media feature, complete the following actions.</span></span>  

1.  <span data-ttu-id="16ced-194">Откройте [командное меню.][DevtoolsCommandMenuIndex]</span><span class="sxs-lookup"><span data-stu-id="16ced-194">Open the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
1.  <span data-ttu-id="16ced-195">Введите `Rendering`.</span><span class="sxs-lookup"><span data-stu-id="16ced-195">Type `Rendering`.</span></span>  
1.  <span data-ttu-id="16ced-196">Запустите **команду отрисовки отображения.**</span><span class="sxs-lookup"><span data-stu-id="16ced-196">Run the **Show Rendering** command.</span></span>  
1.  <span data-ttu-id="16ced-197">Перейдите **к эмулировать цветовую гамму CSS-мультимедиа** и выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="16ced-197">Navigate to **Emulate CSS media feature color-gamut** and choose an option.</span></span>  

<span data-ttu-id="16ced-198">Чтобы узнать больше об этой `color-gamut` функции, перейдите к [качеству отображения цвета: функция "цветовая гамма".][CsswgDraftsMediaqueries4ColorGamut]</span><span class="sxs-lookup"><span data-stu-id="16ced-198">To learn more about the `color-gamut` feature, navigate to [Color Display Quality: the 'color-gamut' feature][CsswgDraftsMediaqueries4ColorGamut].</span></span>  <span data-ttu-id="16ced-199">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1073887][CR1073887].</span><span class="sxs-lookup"><span data-stu-id="16ced-199">To review the history of this feature in the Chromium open-source project, navigate to Issue [1073887][CR1073887].</span></span>  

:::image type="complex" source="../../media/2021/02/rendering-css-color-gamut.msft.png" alt-text="Эмулировать функцию CSS цветовой гаммы мультимедиа" lightbox="../../media/2021/02/rendering-css-color-gamut.msft.png":::
   <span data-ttu-id="16ced-201">Эмулировать функцию CSS цветовой гаммы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="16ced-201">Emulate the CSS color-gamut media feature</span></span>  
:::image-end:::  

### <a name="improved-progressive-web-apps-tooling"></a><span data-ttu-id="16ced-202">Улучшенная прогрессивная программа веб-приложений</span><span class="sxs-lookup"><span data-stu-id="16ced-202">Improved Progressive Web Apps tooling</span></span>  

#### <a name="pwa-installability-warning-in-the-console"></a><span data-ttu-id="16ced-203">Предупреждение об установке PWA в консоли</span><span class="sxs-lookup"><span data-stu-id="16ced-203">PWA installability warning in the Console</span></span>  

<span data-ttu-id="16ced-204">Консоль **теперь** отображает более подробное предупреждение об установке прогрессивных веб-приложений [(PWA)][ProgressiveWebAppsIndex] со ссылкой на улучшение обнаружения поддержки прогрессивного веб-приложения в [автономном режиме.][ChromeDeveloperBlogImprovedPwaOfflineDetection]</span><span class="sxs-lookup"><span data-stu-id="16ced-204">The **Console** now displays a more detailed [Progressive Web Apps (PWA)][ProgressiveWebAppsIndex] installability warning message with a link to [Improving Progressive Web App offline support detection][ChromeDeveloperBlogImprovedPwaOfflineDetection].</span></span>  

:::image type="complex" source="../../media/2021/02/console-pwa-installability.msft.png" alt-text="Предупреждение об установке PWA в консоли" lightbox="../../media/2021/02/console-pwa-installability.msft.png":::
   <span data-ttu-id="16ced-206">Предупреждение об установке PWA в **консоли**</span><span class="sxs-lookup"><span data-stu-id="16ced-206">PWA installability warning in **Console** tool</span></span>  
:::image-end:::  

#### <a name="pwa-description-length-warning-in-the-manifest-pane"></a><span data-ttu-id="16ced-207">Предупреждение о длине описания PWA в области Манифест</span><span class="sxs-lookup"><span data-stu-id="16ced-207">PWA description length warning in the Manifest pane</span></span>

<span data-ttu-id="16ced-208">Теперь **в области Манифест** отображается предупреждение, если описание манифеста превышает 324 символа.</span><span class="sxs-lookup"><span data-stu-id="16ced-208">The **Manifest** pane now displays a warning message if the manifest description exceeds 324 characters.</span></span>  

:::image type="complex" source="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png" alt-text="Предупреждение об усечении описания PWA" lightbox="../../media/2021/02/application-manifest-errors-and-warnings-truncated.msft.png":::
   <span data-ttu-id="16ced-210">Предупреждение об усечении описания PWA</span><span class="sxs-lookup"><span data-stu-id="16ced-210">PWA description truncate warning</span></span>  
:::image-end:::  

<span data-ttu-id="16ced-211">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпускам [965802,][CR965802] [1146450][CR1146450]и [1169689][CR1169689].</span><span class="sxs-lookup"><span data-stu-id="16ced-211">To review the history of this feature in the Chromium open-source project, navigate to Issues [965802][CR965802], [1146450][CR1146450], and [1169689][CR1169689].</span></span>  

### <a name="new-remote-address-space-column-in-the-network-tool"></a><span data-ttu-id="16ced-212">Новый столбец удаленного пространства адресов в средстве Network</span><span class="sxs-lookup"><span data-stu-id="16ced-212">New Remote Address Space column in the Network tool</span></span>  

<!-- does not work in canary 90.0.813.0 -->  
<span data-ttu-id="16ced-213">В новом **столбце Удаленное пространство** адресов отображается сетевое пространство IP-адресов каждого сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="16ced-213">The new **Remote Address Space** column displays the network IP address space of each network resource.</span></span>  <span data-ttu-id="16ced-214">Чтобы отобразить новый столбец Удаленное пространство адресов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="16ced-214">To display the new Remote Address Space column, complete the following actions.</span></span>  

1.  <span data-ttu-id="16ced-215">Перейдите к **средству Network.**</span><span class="sxs-lookup"><span data-stu-id="16ced-215">Navigate to the **Network** tool.</span></span>  
1.  <span data-ttu-id="16ced-216">В таблице Запросы наведите курсор на строку загона и откройте контекстное меню \(правой кнопкой мыши\).</span><span class="sxs-lookup"><span data-stu-id="16ced-216">In the Requests table, hover on the header row, and open the contextual menu \(right-click\).</span></span>  <span data-ttu-id="16ced-217">Чтобы узнать, как добавлять или удалять столбцы из таблицы Запросы, перейдите по добавлению [или удалению столбцов.][DevtoolsNetworkReferenceAddRemoveColumns]</span><span class="sxs-lookup"><span data-stu-id="16ced-217">To learn how to add or remove columns from the Requests table, navigate to [Add or remove columns][DevtoolsNetworkReferenceAddRemoveColumns].</span></span>  
1.  <span data-ttu-id="16ced-218">Выберите **удаленное пространство адресов.**</span><span class="sxs-lookup"><span data-stu-id="16ced-218">Choose **Remote Address Space**.</span></span>  
    
<span data-ttu-id="16ced-219">В таблице Запросы теперь отображается новый столбец с заготвом с именем **Удаленное пространство адресов.**</span><span class="sxs-lookup"><span data-stu-id="16ced-219">The Requests table now displays a new column with the header named **Remote Address Space**.</span></span>  <span data-ttu-id="16ced-220">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1128885][CR1128885].</span><span class="sxs-lookup"><span data-stu-id="16ced-220">To review the history of this feature in the Chromium open-source project, navigate to Issue [1128885][CR1128885].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png" alt-text="В контекстной меню выберите удаленное пространство адресов" lightbox="../../media/2021/02/network-requests-contextual-menu-remote-address-space.msft.png":::
         <span data-ttu-id="16ced-222">В контекстной меню выберите удаленное пространство **адресов**</span><span class="sxs-lookup"><span data-stu-id="16ced-222">In the contextual menu, choose the **Remote Address Space**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/network-requests-remote-address-space.msft.png" alt-text="В таблице Запросы теперь отображается столбец Удаленное пространство адресов" lightbox="../../media/2021/02/network-requests-remote-address-space.msft.png":::
         <span data-ttu-id="16ced-224">В таблице Запросы теперь отображается столбец **Удаленное пространство адресов**</span><span class="sxs-lookup"><span data-stu-id="16ced-224">The Requests table now displays the **Remote Address Space** column</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="display-allowed-and-disallowed-features-in-the-frame-details-view"></a><span data-ttu-id="16ced-225">Отображение разрешенных и отложенных функций в представлении подробностей Frame</span><span class="sxs-lookup"><span data-stu-id="16ced-225">Display allowed and disallowed features in the Frame details view</span></span>  

<span data-ttu-id="16ced-226">Представление сведений о кадре теперь отображает список разрешенных и запрещенных функций браузера, контролируемых [политикой разрешений.][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]</span><span class="sxs-lookup"><span data-stu-id="16ced-226">The Frame details view now displays a list of allowed and disallowed browser features controlled by the [Permissions Policy][GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer].</span></span>  <span data-ttu-id="16ced-227">Политика разрешений — это API веб-платформы, который позволяет \(или blocks\) веб-страницу использовать функции браузера в отдельном кадре или в iframes, которые он встраивал.</span><span class="sxs-lookup"><span data-stu-id="16ced-227">Permissions Policy is a web platform API that allows \(or blocks\) a webpage the use of browser features in an individual frame or in iframes that it embeds.</span></span>  <span data-ttu-id="16ced-228">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1158827][CR1158827].</span><span class="sxs-lookup"><span data-stu-id="16ced-228">To review the history of this feature in the Chromium open-source project, navigate to Issue [1158827][CR1158827].</span></span>  

:::image type="complex" source="../../media/2021/02/application-frames-permissions-policy.msft.png" alt-text="Разрешенные и отостановимые функции на основе политики разрешений" lightbox="../../media/2021/02/application-frames-permissions-policy.msft.png":::
   <span data-ttu-id="16ced-230">Разрешенные и отостановимые функции на основе политики разрешений</span><span class="sxs-lookup"><span data-stu-id="16ced-230">Allowed and disallowed features based on the Permission Policy</span></span>  
:::image-end:::  

### <a name="new-sameparty-column-in-the-cookies-pane"></a><span data-ttu-id="16ced-231">Новый столбец SameParty в области cookies</span><span class="sxs-lookup"><span data-stu-id="16ced-231">New SameParty column in the Cookies pane</span></span>  

<span data-ttu-id="16ced-232">В **области Cookies** в **инструменте Application** теперь отображается атрибут для каждого файла `SameParty` cookie.</span><span class="sxs-lookup"><span data-stu-id="16ced-232">The **Cookies** pane in the **Application** tool now displays the `SameParty` attribute for each cookie.</span></span>  <span data-ttu-id="16ced-233">Атрибут — это новый атрибут boolean, который указывает, включено ли cookie в запросы на истоки тех же `SameParty` [первопартийных наборов.][GithubPrivacycgFirstPartySets]</span><span class="sxs-lookup"><span data-stu-id="16ced-233">The `SameParty` attribute is a new boolean attribute to indicate whether a cookie is included in requests to origins of the same [First-Party Sets][GithubPrivacycgFirstPartySets].</span></span>  <span data-ttu-id="16ced-234">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1161427][CR1161427].</span><span class="sxs-lookup"><span data-stu-id="16ced-234">To review the history of this feature in the Chromium open-source project, navigate to Issue [1161427][CR1161427].</span></span>  

:::image type="complex" source="../../media/2021/02/application-storage-cookies-sameparty.msft.png" alt-text="Столбец SameParty в области Cookies" lightbox="../../media/2021/02/application-storage-cookies-sameparty.msft.png":::
   <span data-ttu-id="16ced-236">**Столбец SameParty** в **области Cookies**</span><span class="sxs-lookup"><span data-stu-id="16ced-236">**SameParty** column in the **Cookies** pane</span></span>  
:::image-end:::  

### <a name="fndisplayname-property-in-the-console-tool-is-now-deprecated"></a><span data-ttu-id="16ced-237">Свойство fn.displayName в средстве Консоли теперь отстает от</span><span class="sxs-lookup"><span data-stu-id="16ced-237">fn.displayName property in the Console tool is now deprecated</span></span>  

<span data-ttu-id="16ced-238">Ранее свойство позволяло управлять отладкой имен для функций, отображаемой в `fn.displayName` `error.stack` и в следах стека DevTools.</span><span class="sxs-lookup"><span data-stu-id="16ced-238">Previously, the `fn.displayName` property allowed you to control debug names for functions to display in `error.stack` and in DevTools stack traces.</span></span>  <span data-ttu-id="16ced-239">Начиная с microsoft Edge версии 90, свойство теперь отстает `fn.displayName` и заменяется `fn.name` свойством.</span><span class="sxs-lookup"><span data-stu-id="16ced-239">Starting in Microsoft Edge version 90, the `fn.displayName` property is now deprecated, and replaced by the `fn.name` property.</span></span>  <span data-ttu-id="16ced-240">Для определения `Object.defineProperty` свойства используйте стандартный `fn.name` метод.</span><span class="sxs-lookup"><span data-stu-id="16ced-240">Use the standard `Object.defineProperty` method to define the `fn.name` property.</span></span>  <span data-ttu-id="16ced-241">Чтобы узнать больше, `fn.name` перейдите к [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span><span class="sxs-lookup"><span data-stu-id="16ced-241">To learn more about `fn.name`, navigate to [Function.name][MdnJavascriptReferenceGlobalObjectsFunctionName].</span></span>  <span data-ttu-id="16ced-242">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [1177685][CR1177685].</span><span class="sxs-lookup"><span data-stu-id="16ced-242">To review the history of this feature in the Chromium open-source project, navigate to Issue [1177685][CR1177685].</span></span>  

:::image type="complex" source="../../media/2021/02/console-display-name-name.msft.png" alt-text="Пример свойства fn.name для управления отлагиванием имен для функций" lightbox="../../media/2021/02/console-display-name-name.msft.png":::
   <span data-ttu-id="16ced-244">Пример свойства `fn.name` для управления отлагиванием имен для функций</span><span class="sxs-lookup"><span data-stu-id="16ced-244">An example of the `fn.name` property to control debug names for functions</span></span>  
:::image-end:::  

### <a name="full-accessibility-tree-view-in-the-elements-tool"></a><span data-ttu-id="16ced-245">Полное представление дерева доступности в средстве Elements</span><span class="sxs-lookup"><span data-stu-id="16ced-245">Full accessibility tree view in the Elements tool</span></span>  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

<span data-ttu-id="16ced-246">Этот эксперимент предоставляет полное представление дерева **доступности** в **средстве Elements.**</span><span class="sxs-lookup"><span data-stu-id="16ced-246">This experiment provides a **full accessibility tree view** in the **Elements** tool.</span></span>  <span data-ttu-id="16ced-247">В [области доступности][DevtoolsAccessibilityReferenceTheAccessibilityPane] обеспечивается частичное представление дерева доступности, которое отображает прямую цепочку предка от корневого узла до проверенного узла.</span><span class="sxs-lookup"><span data-stu-id="16ced-247">The [Accessibility][DevtoolsAccessibilityReferenceTheAccessibilityPane] pane provides a partial accessibility tree view, that displays the direct ancestor chain from the root node to the inspected node.</span></span>  
<span data-ttu-id="16ced-248">После включения этого эксперимента и перезагрузки DevTools выберите одну из следующих кнопок, чтобы переключить дисплей в инструменте Elements для всех элементов на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="16ced-248">After you turn on this experiment and reload the DevTools, choose one of the following buttons to switch the display in the Elements tool for all elements on the webpage.</span></span>  

*   <span data-ttu-id="16ced-249">Чтобы отобразить полное представление дерева доступности, выберите представление **Переключатель дерева доступности.**</span><span class="sxs-lookup"><span data-stu-id="16ced-249">To display the full accessibility tree view , choose the **Switch to Accessibility Tree view**.</span></span>  
*   <span data-ttu-id="16ced-250">Чтобы отобразить представление дерева DOM, выберите представление **Переключатель на дерево DOM.**</span><span class="sxs-lookup"><span data-stu-id="16ced-250">To display the DOM tree view, choose the **Switch to DOM Tree view**.</span></span>  
    
<span data-ttu-id="16ced-251">Чтобы включить эксперимент, перейдите к включив экспериментальные функции и выберите почтовый ящик рядом с включить полное представление дерева доступности в **области Elements.** [][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]</span><span class="sxs-lookup"><span data-stu-id="16ced-251">To turn on the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures] and choose the checkbox next to **Enable full accessibility tree view in Elements pane**.</span></span>  <span data-ttu-id="16ced-252">Чтобы просмотреть историю этой функции в проекте с открытым исходным кодом Chromium, перейдите к выпуску [887173][CR887173].</span><span class="sxs-lookup"><span data-stu-id="16ced-252">To review the history of this feature in the Chromium open-source project, navigate to Issue [887173][CR887173].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png" alt-text="Отображение представления дерева DOM" lightbox="../../media/2021/02/elements-switch-to-accessibility-tree-view.msft.png":::
         <span data-ttu-id="16ced-254">Отображение **представления DOM**</span><span class="sxs-lookup"><span data-stu-id="16ced-254">Display the **DOM view**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png" alt-text="Отображение полного представления дерева доступности" lightbox="../../media/2021/02/elements-switch-to-dom-tree-view.msft.png":::
         <span data-ttu-id="16ced-256">Отображение представления **Дерева полнодоступности**</span><span class="sxs-lookup"><span data-stu-id="16ced-256">Display the **Full Accessibility Tree view**</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="16ced-257">Скачивание Microsoft Edge предварительных каналов</span><span class="sxs-lookup"><span data-stu-id="16ced-257">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="16ced-258">Если вы находитесь на Windows, Linux или macOS, рассмотрите возможность использования каналов предварительного просмотра [Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16ced-258">If you are on Windows, Linux, or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="16ced-259">Предварительные каналы предоставляют доступ к новейшим функциям средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="16ced-259">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="16ced-260">Взаимодействие с командой средств разработчика Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="16ced-260">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  

[DevtoolsAccessibilityReferenceTheAccessibilityPane]: /microsoft-edge/devtools-guide-chromium/accessibility/reference#the-accessibility-pane "Области доступности — справочные | Документы Майкрософт"  
[DevtoolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Запуск команд с командным меню Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsConsoleReferenceFilterByLogLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтр по уровню журнала — консольная справочная | Документы Майкрософт"  
[DevtoolsConsoleReferenceFilterMessages]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-messages "Фильтрация сообщений — справочные | Документы Майкрософт"  
[DevtoolsConsoleReferenceOpenConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console-sidebar "Откройте боковую панель консоли — справочные | Документы Майкрософт"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Параметры — настройка средств разработчика Microsoft Edge | Документация Майкрософт"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Настройка ярлыков клавиатуры в Microsoft Edge DevTools | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexEnablePlusButtonTabMenusToOpenMoreTools]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#enable--button-tab-menus-to-open-more-tools "Включить меню вкладки + кнопки, чтобы открыть дополнительные средства - экспериментальные функции | Документы Майкрософт"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features/index#turn-on-experimental-features "Включаем экспериментальные функции — экспериментальные | Документы Майкрософт"  
[DevtoolsNetworkReferenceAddRemoveColumns]: /microsoft-edge/devtools-guide-chromium/network/reference#add-or-remove-columns "Добавление или удаление столбцов — ссылки на | Документы Майкрософт"  
[DevtoolsNetworkReferenceDisplayInitiatorsDependencies]: /microsoft-edge/devtools-guide-chromium/network/reference#display-initiators-and-dependencies "Отображение инициаторов и зависимостей — справочные | Документы Майкрософт"  

[ProgressiveWebAppsIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения в обзоре Windows | Документы Майкрософт"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Каналы предварительного просмотра Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Обновление расширения вручную — расширение marketplace | Visual Studio Код"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools для Visual Studio кода | Visual Studio Marketplace"  

[ChromeDeveloperBlogImprovedPwaOfflineDetection]: https://developer.chrome.com/blog/improved-pwa-offline-detection "Улучшение обнаружения прогрессивных веб-приложений в автономном режиме | Разработчики Chrome"  

[ChromestatusFeature5354410980933632]: https://www.chromestatus.com/feature/5354410980933632 "запрос мультимедиа с цветовой гаммой | Состояние платформы Chrome"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Ошибки Chromium"  
[CR174309]: https://crbug.com/174309 "Проблема 174309: средства разработчика: разрешение настройки сочетания клавиш | Ошибки Chromium"  
[CR887173]: https://crbug.com/887173 "Выпуск 887173: DevTools: Проверка дерева полной доступности | Ошибки Chromium"  
[CR965802]: https://crbug.com/965802 "Выпуск 965802. Реализация более точного обнаружения автономных возможностей сотрудника службы | Ошибки Chromium"  
[CR1073887]: https://crbug.com/1073887 "Выпуск 1073887: DevTools: @media (цветовая гамма: ...) эмуляция | Ошибки Chromium"  
[CR1128885]: https://crbug.com/1128885 "Выпуск 1128885: поддержка DevTools для corS-RFC1918 | Ошибки Chromium"  
[CR1146450]: https://crbug.com/1146450 "Выпуск 1146450: [Android] Реализация нижнего листа | Ошибки Chromium"  
[CR1158276]: https://crbug.com/1158276 "Выпуск 1158276: невозможно расширить и задать контракт области "Цепочка инициаторов запроса" с помощью клавиш стрелки в разделе "Сеть" в DevTools | Ошибки Chromium"  
[CR1158827]: https://crbug.com/1158827 "Выпуск 1158827: [Политика разрешений] Реализация поддержки devtool политики разрешений | Ошибки Chromium"  
[CR1160637]: https://crbug.com/1160637 "Выпуск 1160637. Фокус на "цепочке инициаторов запроса" рассматривается неполным в разделе "Сеть" окна "Средства разработчика" | Chromium Bugs"  
[CR1161427]: https://crbug.com/1161427 "Выпуск 1161427: &#9730; отладка атрибута cookie SameParty в DevTools | Ошибки Chromium"  
[CR1166710]: https://crbug.com/1166710 "Выпуск 1166710: включить эксперимент по инструментарию flexbox по умолчанию | Ошибки Chromium"  
[CR1169689]: https://crbug.com/1169689 "Выпуск 1169689: нижний лист установки PWA не должен иметь категорий | Ошибки Chromium"  
[CR1175699]: https://crbug.com/1175699 "Выпуск 1175699: редактор Flexbox | Ошибки Chromium"  
[CR1177685]: https://crbug.com/1177685 "Выпуск 1177685: Удаление нестандартной поддержки fn.displayName | Ошибки Chromium"  
[CR1178530]: https://crbug.com/1178530 "Выпуск 1178530: консоль не избегает двойных квотов при печати строк | Ошибки Chromium"  

[CsswgDraftsMediaqueries4ColorGamut]: https://drafts.csswg.org/mediaqueries-4#color-gamut "Качество отображения цвета: функция "цветовая гамма" | Черновики редактора рабочей группы CSS"  

[GithubMicrosoftedgeMsedgeexplainersBlobMainDevtoolsFocusmodeExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DevTools/FocusMode/explainer.md "DevTools: пользовательский интерфейс режима фокуса — MicrosoftEdge/MSEdgeExplainers | GitHub"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft/vscode-edge-devtools | GitHub"  

[GithubPrivacycgFirstPartySets]: https://github.com/privacycg/first-party-sets "Первопартийные наборы | GitHub"  

[GithubW3cWebappsecPermissionsPolicyBlobMainPermissionsPolicyExplainer]: https://github.com/w3c/webappsec-permissions-policy/blob/main/permissions-policy-explainer.md "Объяснятель политики разрешений | GitHub"  

[MdnJavascriptReferenceGlobalObjectsFunctionName]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Function/name "Function.name | MDN"  

> [!NOTE]
> <span data-ttu-id="16ced-300">Некоторые части этой страницы представляют собой измененные материалы, созданные и [предоставленные корпорацией Google][GoogleSitePolicies]. Их использование регулируется условиями, описанными в [лицензии Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="16ced-300">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="16ced-301">Исходная страница находится [здесь](https://developers.google.com/web/updates/2021/02/devtools/index). Ее автор — [Jecelyn Yeen][JecelynYeen] (Джеслин Йен) \(советник по разработке, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="16ced-301">The original page is found [here](https://developers.google.com/web/updates/2021/02/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="16ced-303">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="16ced-303">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
